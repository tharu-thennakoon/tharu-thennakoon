import React from 'react';
import { FaJava, FaPython, FaReact, FaDatabase, FaAngular, FaGithub } from 'react-icons/fa';
import { SiSpringboot, SiJavascript, SiMysql } from 'react-icons/si';

const GithubProfile = () => {
  return (
    <div className="min-h-screen bg-gray-900 text-white p-8 space-y-8 animate-fade-in">
      <header className="text-center space-y-4">
        <h1 className="text-4xl font-bold animate-bounce">
          Hi 👋, I'm Tharushi Thennakoon
        </h1>
        <p className="text-xl text-blue-400 animate-pulse">
          Full Stack Developer
        </p>
        <p className="text-lg text-gray-300">
          Computer Science undergraduate at IIT (University of Westminster)
        </p>
      </header>

      <section className="space-y-6">
        <h2 className="text-2xl font-semibold text-cyan-400">💻 Tech Stack</h2>
        <div className="grid grid-cols-3 md:grid-cols-4 gap-4">
          {[
            { icon: FaJava, name: 'Java', color: 'text-red-500' },
            { icon: FaPython, name: 'Python', color: 'text-yellow-500' },
            { icon: FaReact, name: 'React', color: 'text-blue-400' },
            { icon: SiMysql, name: 'MySQL', color: 'text-orange-400' },
            { icon: SiSpringboot, name: 'Spring Boot', color: 'text-green-500' },
            { icon: SiJavascript, name: 'JavaScript', color: 'text-yellow-300' },
            { icon: FaAngular, name: 'Angular', color: 'text-red-600' }
          ].map((tech, index) => (
            <div 
              key={tech.name}
              className="flex flex-col items-center p-4 bg-gray-800 rounded-lg transform hover:scale-105 transition-transform duration-300"
              style={{ animationDelay: `${index * 100}ms` }}
            >
              <tech.icon className={`text-4xl ${tech.color}`} />
              <span className="mt-2 text-sm">{tech.name}</span>
            </div>
          ))}
        </div>
      </section>

      <section className="space-y-6">
        <h2 className="text-2xl font-semibold text-cyan-400">📊 GitHub Stats</h2>
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div className="bg-gray-800 p-6 rounded-lg animate-fade-in">
            <h3 className="text-xl mb-4">Activity</h3>
            <div className="space-y-2">
              <div className="flex justify-between">
                <span>Total Repositories</span>
                <span className="text-green-400">20</span>
              </div>
              <div className="flex justify-between">
                <span>Stars Earned</span>
                <span className="text-yellow-400">15</span>
              </div>
              <div className="flex justify-between">
                <span>Pull Requests</span>
                <span className="text-purple-400">10</span>
              </div>
            </div>
          </div>
          <div className="bg-gray-800 p-6 rounded-lg animate-fade-in">
            <h3 className="text-xl mb-4">Contributions</h3>
            <div className="h-40 flex items-center justify-center">
              <div className="relative w-32 h-32">
                <div className="absolute inset-0 border-4 border-blue-500 rounded-full animate-ping"></div>
                <div className="absolute inset-0 border-4 border-blue-500 rounded-full"></div>
                <div className="absolute inset-0 flex items-center justify-center">
                  <span className="text-2xl font-bold">500+</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  );
};

export default GithubProfile;
